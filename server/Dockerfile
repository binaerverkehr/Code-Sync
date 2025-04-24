FROM node:18-alpine AS runner

WORKDIR /app

# Kopiere gebaute Artefakte und node_modules
COPY --from=builder /build/dist dist/
COPY --from=builder /build/public public/
COPY --from=builder /build/node_modules ./node_modules
COPY --from=builder /build/package*.json .

EXPOSE 3000

CMD ["npm", "run", "start"]
