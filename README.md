# Ariyana IMs — private encrypted deployments
- `src/` holds the plain memoranda (repo must stay PRIVATE).
- On every push to `main`, GitHub Actions encrypts each file (StatiCrypt, AES-256)
  using the repository secrets PW_BASE / PW_1B / PW_NOFLOW and force-publishes the
  ciphertext to the `deploy` branch (base/ 1b/ noflow/).
- Vercel projects build from the `deploy` branch, one root directory each.
- Never commit passwords; never link the slug domains anywhere public.
